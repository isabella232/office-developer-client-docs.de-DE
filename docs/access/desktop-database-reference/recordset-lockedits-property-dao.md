---
title: Recordset.LockEdits-Eigenschaft (DAO)
TOCTitle: LockEdits Property
ms:assetid: baa11b24-a330-eaa4-bd03-b8b9739d209e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822514(v=office.15)
ms:contentKeyID: 48547379
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052877
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 54f91dea98f4f47057eb673a0fae08c8ac2b6f1c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707710"
---
# <a name="recordsetlockedits-property-dao"></a><span data-ttu-id="bd80b-102">Recordset.LockEdits-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="bd80b-102">Recordset.LockEdits property (DAO)</span></span>

<span data-ttu-id="bd80b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bd80b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bd80b-104">Legt einen Wert fest, der den Typ der Sperreangibt, die während der Bearbeitung wirksam ist, oder gibt diesen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="bd80b-104">Sets or returns a value indicating the type of locking that is in effect while editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd80b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd80b-105">Syntax</span></span>

<span data-ttu-id="bd80b-106">*Ausdruck* . LockEdits</span><span class="sxs-lookup"><span data-stu-id="bd80b-106">*expression* .LockEdits</span></span>

<span data-ttu-id="bd80b-107">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="bd80b-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd80b-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd80b-108">Remarks</span></span>

<span data-ttu-id="bd80b-109">Die Einstellung oder der Rückgabewert gibt den Sperrentyp an, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="bd80b-109">The setting or return value indicates the type of locking, as specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bd80b-110">Wert</span><span class="sxs-lookup"><span data-stu-id="bd80b-110">Value</span></span></p></th>
<th><p><span data-ttu-id="bd80b-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bd80b-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd80b-112">True</span><span class="sxs-lookup"><span data-stu-id="bd80b-112">True</span></span></p></td>
<td><p><span data-ttu-id="bd80b-p101">Standardwert. Eine pessimistische Sperre wird verwendet. Die Seite mit dem aktuell bearbeiteten Datensatz wird gesperrt, sobald Sie die Edit-Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bd80b-p101">Default. Pessimistic locking is in effect. The page containing the record you're editing is locked as soon as you call the Edit method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd80b-116">False</span><span class="sxs-lookup"><span data-stu-id="bd80b-116">False</span></span></p></td>
<td><p><span data-ttu-id="bd80b-117">Parallelität ist für die Bearbeitung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bd80b-117">Optimistic locking is in effect for editing.</span></span> <span data-ttu-id="bd80b-118">Die Seite, die den Datensatz enthält, ist nicht gesperrt, bis die Update-Methode ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bd80b-118">The page containing the record is not locked until the Update method is executed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bd80b-119">Die **LockEdits**-Eigenschaft kann für aktualisierbare **[Recordset](recordset-object-dao.md)** -Objekte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bd80b-119">You can use the **LockEdits** property with updatable **[Recordset](recordset-object-dao.md)** objects.</span></span>

<span data-ttu-id="bd80b-p103">Wenn eine Seite gesperrt ist, kann kein anderer Benutzer Datensätze auf der betreffenden Seite bearbeiten. Wenn Sie für **LockEdits** den Wert **True** festlegen und ein anderer Benutzer die Seite bereits gesperrt hat, tritt ein Fehler auf, wenn Sie die **Edit**-Methode verwenden. Andere Benutzer können Daten aus gesperrten Seiten einlesen.</span><span class="sxs-lookup"><span data-stu-id="bd80b-p103">If a page is locked, no other user can edit records on the same page. If you set **LockEdits** to **True** and another user already has the page locked, an error occurs when you use the **Edit** method. Other users can read data from locked pages.</span></span>

<span data-ttu-id="bd80b-p104">Wenn Sie für die **LockEdits**-Eigenschaft den Wert **False** festlegen und zu einem späteren Zeitpunkt die **Update**-Methode verwenden, während ein anderer Benutzer die Seite gesperrt hat, tritt ein Fehler auf. Mit der **[Move](recordset-move-method-dao.md)** -Methode mit dem Argument 0 können Sie feststellen, welche Änderungen andere Benutzer an Ihrem Datensatz vorgenommen haben. Bei diesem Vorgang gehen jedoch Ihre Änderungen verloren.</span><span class="sxs-lookup"><span data-stu-id="bd80b-p104">If you set the **LockEdits** property to **False** and later use the **Update** method while another user has the page locked, an error occurs. To see the changes made to your record by another user, use the **[Move](recordset-move-method-dao.md)** method with 0 as the argument; however, if you do this, you will lose your changes.</span></span>

<span data-ttu-id="bd80b-p105">Wenn Sie ODBC-Datenquellen verwenden, die mit der Microsoft Access-Datenbank-Engine verbunden sind, ist für die **LockEdits**-Eigenschaft immer **False** bzw. die optimistische Sperre festgelegt. Die Microsoft Access-Datenbank-Engine hat keine Kontrolle über die von externen Datenbankservern verwendeten Sperrmechanismen.</span><span class="sxs-lookup"><span data-stu-id="bd80b-p105">When working with Microsoft Access database engine-connected ODBC data sources, the **LockEdits** property is always set to **False**, or optimistic locking. The Microsoft Access database engine has no control over the locking mechanisms used in external database servers.</span></span>

> [!NOTE]
> <span data-ttu-id="bd80b-127">Sie können den Wert der **LockEdits** voreinstellen, wenn Sie das **Recordset-Objekt** zunächst öffnen, indem Sie das Argument Sperren der **[OpenRecordset](connection-openrecordset-method-dao.md)** -Methode festlegen.</span><span class="sxs-lookup"><span data-stu-id="bd80b-127">You can preset the value of **LockEdits** when you first open the **Recordset** by setting the lockedits argument of the **[OpenRecordset](connection-openrecordset-method-dao.md)** method.</span></span> <span data-ttu-id="bd80b-128">Festlegen des Arguments Lockedits auf **DbPessimistic** **LockEdits** -Eigenschaft auf **True**festgelegt wird, und Einstellung Lockedits auf einen anderen Wert wird die **LockEdits** -Eigenschaft auf **False**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bd80b-128">Setting the lockedits argument to **dbPessimistic** will set the **LockEdits** property to **True**, and setting lockedits to any other value will set the **LockEdits** property to **False**.</span></span>

## <a name="example"></a><span data-ttu-id="bd80b-129">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bd80b-129">Example</span></span>

<span data-ttu-id="bd80b-p107">In diesem Beispiel wird die pessimistische Sperre veranschaulicht, indem die LockEdits-Eigenschaft auf True festgelegt wird. Dann wird die optimistische Sperre verwendet, indem die LockEdits-Eigenschaft auf False festgelegt wird. Außerdem wird gezeigt, welche Art von Fehlerbehandlung in einer Mehrbenutzerdatenbank-Umgebung erforderlich ist, um ein Feld zu ändern. Damit diese Prozedur ausgeführt werden kann, sind die Funktionen PessimisticLock und OptimisticLock erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bd80b-p107">This example demonstrates pessimistic locking by setting the **LockEdits** property to **True**, and then demonstrates optimistic locking by setting the **LockEdits** property to False. It also demonstrates what kind of error handling is required in a multiuser database environment in order to modify a field. The PessimisticLock and OptimisticLock functions are required for this procedure to run.</span></span>

```vb
    Sub LockEditsX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCustomers As Recordset 
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
     
    Function PessimisticLock(rstTemp As Recordset, _ 
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
