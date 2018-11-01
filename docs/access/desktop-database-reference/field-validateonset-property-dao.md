---
title: Field.ValidateOnSet Property (DAO)
TOCTitle: ValidateOnSet Property
ms:assetid: 00245a8a-a78f-b0a8-3eb3-11dd27873984
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844720(v=office.15)
ms:contentKeyID: 48542898
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052929
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9a7f89277b51ef0edb5603c4482d4547201673fb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884773"
---
# <a name="fieldvalidateonset-property-dao"></a><span data-ttu-id="78d2e-102">Field.ValidateOnSet Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="78d2e-102">Field.ValidateOnSet Property (DAO)</span></span>


<span data-ttu-id="78d2e-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="78d2e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="78d2e-104">Legt einen Wert fest, der angibt, ob der Wert eines **[Field](field-object-dao.md)** -Objekts sofort der Gültigkeitsprüfung unterzogen wird, wenn die **[Value](field-value-property-dao.md)** -Eigenschaft des Objekts festgelegt wird, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="78d2e-104">Sets or returns a value that specifies whether or not the value of a **[Field](field-object-dao.md)** object is immediately validated when the object's **[Value](field-value-property-dao.md)** property is set (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="78d2e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="78d2e-105">Syntax</span></span>

<span data-ttu-id="78d2e-106">*Ausdruck* . ValidateOnSet</span><span class="sxs-lookup"><span data-stu-id="78d2e-106">*expression* .ValidateOnSet</span></span>

<span data-ttu-id="78d2e-107">*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="78d2e-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="78d2e-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78d2e-108">Remarks</span></span>

<span data-ttu-id="78d2e-109">Nur **Field**-Objekte in **[Recordset](recordset-object-dao.md)** -Objekten unterstützen die **ValidateOnSet**-Eigenschaft mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="78d2e-109">Only **Field** objects in **[Recordset](recordset-object-dao.md)** objects support the **ValidateOnSet** property as read/write.</span></span>

<span data-ttu-id="78d2e-110">**ValidateOnSet** -Eigenschaft auf **True** festlegen kann in einer Situation nützlich sein, wenn ein Benutzer Datensätze eingibt, die erhebliche Memodaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="78d2e-110">Setting the **ValidateOnSet** property to **True** can be useful in a situation when a user is entering records that include substantial Memo data.</span></span> <span data-ttu-id="78d2e-111">Warten, bis das **[Update](recordset-update-method-dao.md)** aufrufen, um die Daten überprüfen kann dazu führen unnötige Zeitaufwand für das Schreiben der langen Memo-Daten in der Datenbank, wenn es stellt sich darauf hin, dass die Daten ungültig waren, da eine Überprüfungsregel in einem anderen Feld unterbrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="78d2e-111">Waiting until the **[Update](recordset-update-method-dao.md)** call to validate the data can result in unnecessary time spent writing the lengthy Memo data to the database if it turns out that the data was invalid anyway because a validation rule was broken in another field.</span></span>

## <a name="example"></a><span data-ttu-id="78d2e-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="78d2e-112">Example</span></span>

<span data-ttu-id="78d2e-p102">Diese Beispiel veranschaulicht mit der ValidateOnSet-Eigenschaft, wie Fehler bei der Dateneingabe abgefangen werden können. Zum Ausführen dieser Prozedur ist die ValidateData-Funktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="78d2e-p102">This example uses the **ValidateOnSet** property to demonstrate how one might trap for errors during data entry. The ValidateData function is required for this procedure to run.</span></span>

```vb
    Sub ValidateOnSetX() 
     
     Dim dbsNorthwind As Database 
     Dim fldDays As Field 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create and append a new Field object to the Fields 
     ' collection of the Employees table. 
     Set fldDays = _ 
     dbsNorthwind.TableDefs!Employees.CreateField( _ 
     "DaysOfVacation", dbInteger, 2) 
     fldDays.ValidationRule = "BETWEEN 1 AND 20" 
     fldDays.ValidationText = _ 
     "Number must be between 1 and 20!" 
     dbsNorthwind.TableDefs!Employees.Fields.Append fldDays 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     
     Do While True 
     ' Add new record. 
     .AddNew 
     
     ' Get user input for three fields. Verify that the 
     ' data do not violate the validation rules for any 
     ' of the fields. 
     If ValidateData(!FirstName, _ 
     "Enter first name.") = False Then Exit Do 
     If ValidateData(!LastName, _ 
     "Enter last name.") = False Then Exit Do 
     If ValidateData(!DaysOfVacation, _ 
     "Enter days of vacation.") = False Then Exit Do 
     
     .Update 
     .Bookmark = .LastModified 
     Debug.Print !FirstName & " " & !LastName & _ 
     " - " & "DaysOfVacation = " & !DaysOfVacation 
     
     ' Delete new record because this is a demonstration. 
     .Delete 
     Exit Do 
     Loop 
     
     ' Cancel AddNew method if any of the validation rules 
     ' were broken. 
     If .EditMode <> dbEditNone Then .CancelUpdate 
     .Close 
     End With 
     
     ' Delete new field because this is a demonstration. 
     dbsNorthwind.TableDefs!Employees.Fields.Delete _ 
     fldDays.Name 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function ValidateData(fldTemp As Field, _ 
     strMessage As String) As Boolean 
     
     Dim strInput As String 
     Dim errLoop As Error 
     
     ValidateData = True 
     ' ValidateOnSet is only read/write for Field objects in 
     ' Recordset objects. 
     fldTemp.ValidateOnSet = True 
     
     Do While True 
     strInput = InputBox(strMessage) 
     If strInput = "" Then Exit Do 
     ' Trap for errors when setting the Field value. 
     On Error GoTo Err_Data 
     If fldTemp.Type = dbInteger Then 
     fldTemp = Val(strInput) 
     Else 
     fldTemp = strInput 
     End If 
     On Error GoTo 0 
     If Not IsNull(fldTemp) Then Exit Do 
     Loop 
     
     If strInput = "" Then ValidateData = False 
     
     Exit Function 
     
    Err_Data: 
     
     If DBEngine.Errors.Count > 0 Then 
     ' Enumerate the Errors collection. The description 
     ' property of the last Error object will be set to 
     ' the ValidationText property of the relevant 
     ' field. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     End If 
     
     Resume Next 
     
    End Function
```
