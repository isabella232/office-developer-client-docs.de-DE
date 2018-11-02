---
title: Recordset2.LockEdits-Eigenschaft (DAO)
TOCTitle: LockEdits Property
ms:assetid: 77055f44-f8e9-ac64-ecc3-144ddb4a4558
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196045(v=office.15)
ms:contentKeyID: 48545716
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f93924c579dc32e0841177eeb1068df64e12ab9b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931085"
---
# <a name="recordset2lockedits-property-dao"></a>Recordset2.LockEdits-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

Legt einen Wert fest, der den Typ der Sperreangibt, die während der Bearbeitung wirksam ist, oder gibt diesen Wert zurück.

## <a name="syntax"></a>Syntax

*Ausdruck* . LockEdits

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die Einstellung oder der Rückgabewert gibt den Sperrentyp an, wie in der folgenden Tabelle dargestellt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Wert</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>True</p></td>
<td><p>Standardwert. Eine pessimistische Sperre wird verwendet. Die Seite mit dem aktuell bearbeiteten Datensatz wird gesperrt, sobald Sie die Edit-Methode aufrufen.</p></td>
</tr>
<tr class="even">
<td><p>False</p></td>
<td><p>Parallelität ist für die Bearbeitung aktiviert. Die Seite, die den Datensatz enthält, ist nicht gesperrt, bis die Update-Methode ausgeführt wird.</p></td>
</tr>
</tbody>
</table>


Die **LockEdits**-Eigenschaft kann für aktualisierbare **[Recordset](recordset-object-dao.md)** -Objekte verwendet werden.

Wenn eine Seite gesperrt ist, kann kein anderer Benutzer Datensätze auf der betreffenden Seite bearbeiten. Wenn Sie für **LockEdits** den Wert **True** festlegen und ein anderer Benutzer die Seite bereits gesperrt hat, tritt ein Fehler auf, wenn Sie die **Edit**-Methode verwenden. Andere Benutzer können Daten aus gesperrten Seiten einlesen.

Wenn Sie für die **LockEdits**-Eigenschaft den Wert **False** festlegen und zu einem späteren Zeitpunkt die **Update**-Methode verwenden, während ein anderer Benutzer die Seite gesperrt hat, tritt ein Fehler auf. Mit der **[Move](recordset2-move-method-dao.md)** -Methode mit dem Argument 0 können Sie feststellen, welche Änderungen andere Benutzer an Ihrem Datensatz vorgenommen haben. Bei diesem Vorgang gehen jedoch Ihre Änderungen verloren.

Wenn Sie ODBC-Datenquellen verwenden, die mit der Microsoft Access-Datenbank-Engine verbunden sind, ist für die **LockEdits**-Eigenschaft immer **False** bzw. die optimistische Sperre festgelegt. Die Microsoft Access-Datenbank-Engine hat keine Kontrolle über die von externen Datenbankservern verwendeten Sperrmechanismen.


> [!NOTE]
> <P>Sie können den Wert der <STRONG>LockEdits</STRONG> voreinstellen, wenn Sie das <STRONG>Recordset-Objekt</STRONG> zunächst öffnen, indem Sie das Argument Sperren der <STRONG><A href="connection-openrecordset-method-dao.md">OpenRecordset</A></STRONG> -Methode festlegen. Festlegen des Arguments Lockedits auf <STRONG>DbPessimistic</STRONG> <STRONG>LockEdits</STRONG> -Eigenschaft auf <STRONG>True</STRONG>festgelegt wird, und Einstellung Lockedits auf einen anderen Wert wird die <STRONG>LockEdits</STRONG> -Eigenschaft auf <STRONG>False</STRONG>festgelegt.</P>



## <a name="example"></a>Beispiel

In diesem Beispiel wird die pessimistische Sperre veranschaulicht, indem die LockEdits-Eigenschaft auf True festgelegt wird. Dann wird die optimistische Sperre verwendet, indem die LockEdits-Eigenschaft auf False festgelegt wird. Außerdem wird gezeigt, welche Art von Fehlerbehandlung in einer Mehrbenutzerdatenbank-Umgebung erforderlich ist, um ein Feld zu ändern. Damit diese Prozedur ausgeführt werden kann, sind die Funktionen PessimisticLock und OptimisticLock erforderlich.

```vb
    Sub LockEditsX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCustomers As Recordset2 
     Dim strOldName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCustomers = _ 
     dbsNorthwind.OpenRecordset("Customers", _ 
     dbOpenDynaset) 
     
     With rstCustomers 
     ' Store original data. 
     strOldName = !CompanyName 
     
     If MsgBox("Pessimistic locking demonstration...", _ 
     vbOKCancel) = vbOK Then 
     
     ' Attempt to modify data with pessimistic locking 
     ' in effect. 
     If PessimisticLock(rstCustomers, !CompanyName, _ 
     "Acme Foods") Then 
     MsgBox "Record successfully edited." 
     
     ' Restore original data... 
     .Edit 
     !CompanyName = strOldName 
     .Update 
     End If 
     
     End If 
     
     If MsgBox("Optimistic locking demonstration...", _ 
     vbOKCancel) = vbOK Then 
     
     ' Attempt to modify data with optimistic locking 
     ' in effect. 
     If OptimisticLock(rstCustomers, !CompanyName, _ 
     "Acme Foods") Then 
     MsgBox "Record successfully edited." 
     
     ' Restore original data... 
     .Edit 
     !CompanyName = strOldName 
     .Update 
     End If 
     
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function PessimisticLock(rstTemp As Recordset2, _ 
     fldTemp As Field, strNew As String) As Boolean 
     
     dim ErrLoop as Error 
     
     PessimisticLock = True 
     
     With rstTemp 
     .LockEdits = True 
     
     ' When you set LockEdits to True, you trap for errors 
     ' when you call the Edit method. 
     On Error GoTo Err_Lock 
     .Edit 
     On Error GoTo 0 
     
     ' If the Edit is still in progress, then no errors 
     ' were triggered; you may modify the data. 
     If .EditMode = dbEditInProgress Then 
     fldTemp = strNew 
     .Update 
     .Bookmark = .LastModified 
     Else 
     ' Retrieve current record to see changes made by 
     ' other user. 
     .Move 0 
     End If 
     
     End With 
     
     Exit Function 
     
    Err_Lock: 
     
     If DBEngine.Errors.Count > 0 Then 
     ' Enumerate the Errors collection. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     PessimisticLock = False 
     End If 
     
     Resume Next 
     
    End Function 
     
    Function OptimisticLock(rstTemp As Recordset, _ 
     fldTemp As Field, strNew As String) As Boolean 
     
     dim ErrLoop as Error 
     
     OptimisticLock = True 
     
     With rstTemp 
     .LockEdits = False 
     .Edit 
     fldTemp = strNew 
     
     ' When you set LockEdits to False, you trap for errors 
     ' when you call the Update method. 
     On Error GoTo Err_Lock 
     .Update 
     On Error GoTo 0 
     
     ' If there is no Edit in progress, then no errors were 
     ' triggered; you may modify the data. 
     If .EditMode = dbEditNone Then 
     ' Move current record pointer to the most recently 
     ' modified record. 
     .Bookmark = .LastModified 
     Else 
     .CancelUpdate 
     ' Retrieve current record to see changes made by 
     ' other user. 
     .Move 0 
     End If 
     
     End With 
     
     Exit Function 
     
    Err_Lock: 
     
     If DBEngine.Errors.Count > 0 Then 
     ' Enumerate the Errors collection. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     OptimisticLock = False 
     End If 
     
     Resume Next 
     
    End Function
```
