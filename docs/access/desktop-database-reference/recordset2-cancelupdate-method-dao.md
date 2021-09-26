---
title: Recordset2.CancelUpdate-Methode (DAO)
TOCTitle: CancelUpdate Method
ms:assetid: f741dec1-b9a4-506e-74ec-2bc309b0918e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836907(v=office.15)
ms:contentKeyID: 48548761
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4081902037e33b5ed940e44b2b27f4ffd75593e2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631783"
---
# <a name="recordset2cancelupdate-method-dao"></a>Recordset2.CancelUpdate-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Bricht alle ausstehenden Updates für ein **[Recordset](recordset-object-dao.md)**-Objekt ab.

## <a name="syntax"></a>Syntax

*Ausdruck* . CancelUpdate(***UpdateType***)

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
<td><p><em>UpdateType</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Auf einen der <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum-Werte</a></strong> festgelegt.</p><p><strong>HINWEIS:</strong>Die Werte <EM>"dbUpdateRegular"</EM> und <EM>"dbUpdateBatch"</EM> sind nur gültig, wenn die Batchaktualisierung aktiviert ist.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Mit der **CancelUpdate**-Methode können Sie alle ausstehenden Aktualisierungen abbrechen, die aus einer **[Edit](recordset2-edit-method-dao.md)** - oder **[AddNew](recordset2-addnew-method-dao.md)** -Operation stammen. Wenn ein Benutzer z. B. die **Edit**- oder **AddNew**-Methode aufruft, ohne vorher die **Update**-Methode aufgerufen zu haben, werden durch die **CancelUpdate**-Methode alle Änderungen abgebrochen, die nach dem Aufrufen von **Edit** oder **AddNew** vorgenommen wurden.

Überprüfen Sie die **[EditMode](recordset2-editmode-property-dao.md)** -Eigenschaft des **Recordset**-Objekts, um zu ermitteln, ob eine Operation aussteht, die abgebrochen werden kann.

> [!NOTE]
> [!HINWEIS] Die Verwendung der **CancelUpdate**-Methode hat dieselbe Wirkung wie das Verschieben zu einem anderen Datensatz, ohne die **[Update](recordset2-update-method-dao.md)** -Methode zu verwenden. Der einzige Unterschied besteht darin, dass der aktuelle Datensatz nicht geändert wird und dass verschiedene Eigenschaften nicht aktualisiert werden, z. B. **[BOF](recordset2-bof-property-dao.md)** und **[EOF](recordset2-eof-property-dao.md)**.

## <a name="example"></a>Beispiel

Dieses Beispiel zeigt, wie die Methoden **CancelUpdate** und **AddNew** kombiniert werden.

```vb
    Sub CancelUpdateX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset2 
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

